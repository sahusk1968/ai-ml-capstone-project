import random

# --- Utility Functions ---

def generate_random(dim):

    return [random.uniform(0, 1) for _ in range(dim)]

def clamp(values):

    return [min(1, max(0, v)) for v in values]

def tweak(values, step):

    return clamp([v + random.uniform(-step, step) for v in values])

# --- Initial Random Search (Week 1–2) ---

def random_search():

    return {
    
        "f1": generate_random(2),
        
        "f2": generate_random(2),
        
        "f3": generate_random(3),
        
        "f4": generate_random(4),
        
        "f5": generate_random(4),
        
        "f6": generate_random(5),
        
        "f7": generate_random(6),
        
        "f8": generate_random(8),
    }

# --- Local Optimization ---

def local_search(prev, step):

    return {k: tweak(v, step) for k, v in prev.items()}

# --- Guided Directional Search ---

def guided_search(values, direction, step=0.02):

    return clamp([v + step * d for v, d in zip(values, direction)])

# --- Main Strategy Controller ---

def optimization_pipeline(week, prev_best=None):
    
    # Week 1–2: Random exploration
    
    if week in [1, 2]:
    
        return random_search()
    
    # Week 3–4: Local tuning
    
    elif week in [3, 4]:
    
        return local_search(prev_best, step=0.05 if week == 3 else 0.02)
    
    # Week 5: Exploration reset
    
    elif week == 5:
    
        return random_search()
    
    # Week 6–7: Refinement
    
    elif week in [6, 7]:
    
        return local_search(prev_best, step=0.03 if week == 6 else 0.01)
    
    # Week 8–9: Guided tuning
    
    elif week in [8, 9]:
    
        return local_search(prev_best, step=0.02)
    
    # Week 10–11: Fine-tuning (convergence)
    
    elif week in [10, 11]:
    
        return local_search(prev_best, step=0.005)
    
    # Week 12: Slight exploration
    
    elif week == 12:
    
        return local_search(prev_best, step=0.02)
    
    # Week 13: Final refinement
    
    elif week == 13:
    
        return local_search(prev_best, step=0.005)
    
    else:
    
        raise ValueError("Invalid week")

# Example usage

current = random_search()

for week in range(1, 14):

    current = optimization_pipeline(week, current)
    
    print(f"Week {week} inputs:", current)
